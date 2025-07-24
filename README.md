# hello-github
Just doing the ChatGPT guide, nothing to see here
This is my first GitHub respository
This is my first commit!
This change is on the feature-1 branch
import { Button } from '@/components/ui/button';
import { Card, CardContent, CardHeader, CardTitle } from '@/components/ui/card';
import { motion } from 'framer-motion';

export default function MentorshipWebsite() {
  return (
    <div className="bg-gray-50 min-h-screen p-6">
      <header className="text-center py-10">
        <h1 className="text-4xl font-bold mb-3">LeadersLikeMe Mentorship</h1>
        <p className="text-lg text-gray-600">
          Empowering students from less advantaged communities through dedicated mentorship and support.
        </p>
        <Button className="mt-5">Join as Mentor</Button>
      </header>

      <section className="grid md:grid-cols-3 gap-6 my-8">
        {['Personal Growth', 'Academic Support', 'Career Guidance'].map((program) => (
          <motion.div
            key={program}
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6 }}
          >
            <Card className="shadow-lg">
              <CardHeader>
                <CardTitle>{program}</CardTitle>
              </CardHeader>
              <CardContent>
                <p className="text-gray-600">
                  Tailored mentorship programs designed to foster {program.toLowerCase()} and empowerment.
                </p>
              </CardContent>
            </Card>
          </motion.div>
        ))}
      </section>

      <section className="my-12 bg-white shadow rounded-xl p-6">
        <h2 className="text-2xl font-bold text-center mb-4">Our Impact</h2>
        <div className="grid md:grid-cols-2 gap-4">
          <p className="text-gray-600">
            "Thanks to LeadersLikeMe, I've achieved milestones I never thought possible!" – <strong>Maria, High School Senior</strong>
          </p>
          <p className="text-gray-600">
            "My mentor provided crucial guidance and confidence to pursue higher education." – <strong>Jamal, College Student</strong>
          </p>
        </div>
      </section>

      <footer className="text-center py-8">
        <p className="mb-4 text-gray-500">Support our cause and help us reach more students.</p>
        <Button variant="outline">Donate Now</Button>
      </footer>
    </div>
  );
}
